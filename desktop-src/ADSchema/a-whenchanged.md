---
title: When-Changed 屬性
description: 上次變更此物件的日期。 此值不會複寫，而且存在於通用類別目錄中。
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- When-Changed 屬性 AD 架構
- whenChanged 屬性 AD 架構
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844539"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="e5e0e-106">When-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="e5e0e-106">When-Changed attribute</span></span>

<span data-ttu-id="e5e0e-107">上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="e5e0e-107">The date when this object was last changed.</span></span> <span data-ttu-id="e5e0e-108">此值不會複寫，而且存在於通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="e5e0e-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="e5e0e-109">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-109">Entry</span></span> | <span data-ttu-id="e5e0e-110">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="e5e0e-111">CN</span><span class="sxs-lookup"><span data-stu-id="e5e0e-111">CN</span></span>                | <span data-ttu-id="e5e0e-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="e5e0e-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="e5e0e-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e5e0e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e5e0e-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="e5e0e-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="e5e0e-115">大小</span><span class="sxs-lookup"><span data-stu-id="e5e0e-115">Size</span></span>              | <span data-ttu-id="e5e0e-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="e5e0e-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="e5e0e-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e5e0e-117">Update Privilege</span></span>  | <span data-ttu-id="e5e0e-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e5e0e-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="e5e0e-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e5e0e-119">Update Frequency</span></span>  | <span data-ttu-id="e5e0e-120">每次物件變更時。</span><span class="sxs-lookup"><span data-stu-id="e5e0e-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="e5e0e-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-121">Attribute-Id</span></span>      | <span data-ttu-id="e5e0e-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="e5e0e-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="e5e0e-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e5e0e-123">System-Id-Guid</span></span>    | <span data-ttu-id="e5e0e-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e5e0e-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="e5e0e-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e0e-125">Syntax</span></span>            | [<span data-ttu-id="e5e0e-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="e5e0e-127">實作</span><span class="sxs-lookup"><span data-stu-id="e5e0e-127">Implementations</span></span>

-   [<span data-ttu-id="e5e0e-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5e0e-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5e0e-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e5e0e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5e0e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5e0e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5e0e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5e0e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5e0e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e5e0e-136">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-136">Entry</span></span> | <span data-ttu-id="e5e0e-137">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-139">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-140">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-141">System-Only</span></span>            | <span data-ttu-id="e5e0e-142">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-142">True</span></span>                            |
| <span data-ttu-id="e5e0e-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-144">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-144">True</span></span>                            |
| <span data-ttu-id="e5e0e-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-145">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-146">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-146">False</span></span>                           |
| <span data-ttu-id="e5e0e-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-147">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-148">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-148">True</span></span>                            |
| <span data-ttu-id="e5e0e-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-153">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-154">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-155">System-Flags</span></span>           | <span data-ttu-id="e5e0e-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-156">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-157">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5e0e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5e0e-159">Windows Server 2003</span></span>



| <span data-ttu-id="e5e0e-160">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-160">Entry</span></span> | <span data-ttu-id="e5e0e-161">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-163">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-164">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-165">System-Only</span></span>            | <span data-ttu-id="e5e0e-166">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-166">True</span></span>                            |
| <span data-ttu-id="e5e0e-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-167">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-168">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-168">True</span></span>                            |
| <span data-ttu-id="e5e0e-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-169">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-170">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-170">False</span></span>                           |
| <span data-ttu-id="e5e0e-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-171">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-172">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-172">True</span></span>                            |
| <span data-ttu-id="e5e0e-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-177">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-178">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-179">System-Flags</span></span>           | <span data-ttu-id="e5e0e-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-180">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-181">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e5e0e-183">亞當</span><span class="sxs-lookup"><span data-stu-id="e5e0e-183">ADAM</span></span>



| <span data-ttu-id="e5e0e-184">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-184">Entry</span></span> | <span data-ttu-id="e5e0e-185">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-187">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-188">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-189">System-Only</span></span>            | <span data-ttu-id="e5e0e-190">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-190">True</span></span>                            |
| <span data-ttu-id="e5e0e-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-192">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-192">True</span></span>                            |
| <span data-ttu-id="e5e0e-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-193">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-194">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-194">False</span></span>                           |
| <span data-ttu-id="e5e0e-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-195">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-196">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-196">True</span></span>                            |
| <span data-ttu-id="e5e0e-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-201">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-202">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-203">System-Flags</span></span>           | <span data-ttu-id="e5e0e-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-204">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-205">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5e0e-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5e0e-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5e0e-208">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-208">Entry</span></span> | <span data-ttu-id="e5e0e-209">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-211">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-212">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-213">System-Only</span></span>            | <span data-ttu-id="e5e0e-214">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-214">True</span></span>                            |
| <span data-ttu-id="e5e0e-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-215">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-216">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-216">True</span></span>                            |
| <span data-ttu-id="e5e0e-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-217">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-218">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-218">False</span></span>                           |
| <span data-ttu-id="e5e0e-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-219">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-220">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-220">True</span></span>                            |
| <span data-ttu-id="e5e0e-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-225">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-226">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-227">System-Flags</span></span>           | <span data-ttu-id="e5e0e-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-228">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-229">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5e0e-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-231">Windows Server 2008</span></span>



| <span data-ttu-id="e5e0e-232">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-232">Entry</span></span> | <span data-ttu-id="e5e0e-233">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-235">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-236">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-237">System-Only</span></span>            | <span data-ttu-id="e5e0e-238">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-238">True</span></span>                            |
| <span data-ttu-id="e5e0e-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-239">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-240">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-240">True</span></span>                            |
| <span data-ttu-id="e5e0e-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-241">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-242">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-242">False</span></span>                           |
| <span data-ttu-id="e5e0e-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-243">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-244">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-244">True</span></span>                            |
| <span data-ttu-id="e5e0e-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-249">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-250">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-251">System-Flags</span></span>           | <span data-ttu-id="e5e0e-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-252">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-253">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5e0e-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5e0e-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5e0e-256">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-256">Entry</span></span> | <span data-ttu-id="e5e0e-257">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-259">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-260">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-261">System-Only</span></span>            | <span data-ttu-id="e5e0e-262">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-262">True</span></span>                            |
| <span data-ttu-id="e5e0e-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-264">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-264">True</span></span>                            |
| <span data-ttu-id="e5e0e-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-265">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-266">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-266">False</span></span>                           |
| <span data-ttu-id="e5e0e-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-267">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-268">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-268">True</span></span>                            |
| <span data-ttu-id="e5e0e-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-273">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-274">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-275">System-Flags</span></span>           | <span data-ttu-id="e5e0e-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-276">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-277">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5e0e-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5e0e-279">Windows Server 2012</span></span>



| <span data-ttu-id="e5e0e-280">進入</span><span class="sxs-lookup"><span data-stu-id="e5e0e-280">Entry</span></span> | <span data-ttu-id="e5e0e-281">值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e5e0e-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e0e-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e5e0e-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e0e-283">MAPI-Id</span></span>                | <span data-ttu-id="e5e0e-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="e5e0e-284">0x3008</span></span>                          |
| <span data-ttu-id="e5e0e-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e0e-285">System-Only</span></span>            | <span data-ttu-id="e5e0e-286">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-286">True</span></span>                            |
| <span data-ttu-id="e5e0e-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5e0e-287">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e0e-288">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-288">True</span></span>                            |
| <span data-ttu-id="e5e0e-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5e0e-289">Is Indexed</span></span>             | <span data-ttu-id="e5e0e-290">否</span><span class="sxs-lookup"><span data-stu-id="e5e0e-290">False</span></span>                           |
| <span data-ttu-id="e5e0e-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5e0e-291">In Global Catalog</span></span>      | <span data-ttu-id="e5e0e-292">對</span><span class="sxs-lookup"><span data-stu-id="e5e0e-292">True</span></span>                            |
| <span data-ttu-id="e5e0e-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5e0e-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e0e-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5e0e-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e5e0e-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e0e-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e0e-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e5e0e-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-297">Search-Flags</span></span>           | <span data-ttu-id="e5e0e-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0e-298">0x00000000</span></span>                      |
| <span data-ttu-id="e5e0e-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e0e-299">System-Flags</span></span>           | <span data-ttu-id="e5e0e-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e5e0e-300">0x00000013</span></span>                      |
| <span data-ttu-id="e5e0e-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5e0e-301">Classes used in</span></span>        | [<span data-ttu-id="e5e0e-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e5e0e-302">**Top**</span></span>](c-top.md)<br/> |



 

 





