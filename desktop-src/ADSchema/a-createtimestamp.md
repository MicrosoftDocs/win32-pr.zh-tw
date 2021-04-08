---
title: 建立時間戳記屬性
description: 此物件的建立日期。 此值為已複寫。
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- 建立時間戳記屬性 AD 架構
- createTimeStamp 屬性 AD 架構
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687311"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="ac0db-106">建立時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="ac0db-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="ac0db-107">此物件的建立日期。</span><span class="sxs-lookup"><span data-stu-id="ac0db-107">The date when this object was created.</span></span> <span data-ttu-id="ac0db-108">此值為已複寫。</span><span class="sxs-lookup"><span data-stu-id="ac0db-108">This value is replicated.</span></span>



| <span data-ttu-id="ac0db-109">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-109">Entry</span></span> | <span data-ttu-id="ac0db-110">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="ac0db-111">CN</span><span class="sxs-lookup"><span data-stu-id="ac0db-111">CN</span></span>                | <span data-ttu-id="ac0db-112">建立時間戳記</span><span class="sxs-lookup"><span data-stu-id="ac0db-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="ac0db-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ac0db-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ac0db-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ac0db-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="ac0db-115">大小</span><span class="sxs-lookup"><span data-stu-id="ac0db-115">Size</span></span>              | <span data-ttu-id="ac0db-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="ac0db-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="ac0db-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ac0db-117">Update Privilege</span></span>  | <span data-ttu-id="ac0db-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ac0db-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="ac0db-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ac0db-119">Update Frequency</span></span>  | <span data-ttu-id="ac0db-120">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="ac0db-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="ac0db-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-121">Attribute-Id</span></span>      | <span data-ttu-id="ac0db-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="ac0db-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="ac0db-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ac0db-123">System-Id-Guid</span></span>    | <span data-ttu-id="ac0db-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="ac0db-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="ac0db-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac0db-125">Syntax</span></span>            | [<span data-ttu-id="ac0db-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="ac0db-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="ac0db-127">實作</span><span class="sxs-lookup"><span data-stu-id="ac0db-127">Implementations</span></span>

-   [<span data-ttu-id="ac0db-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac0db-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac0db-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac0db-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac0db-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ac0db-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ac0db-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac0db-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac0db-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac0db-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac0db-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac0db-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac0db-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac0db-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac0db-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac0db-135">Windows 2000 Server</span></span>



| <span data-ttu-id="ac0db-136">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-136">Entry</span></span> | <span data-ttu-id="ac0db-137">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-140">System-Only</span></span>            | <span data-ttu-id="ac0db-141">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-141">True</span></span>                            |
| <span data-ttu-id="ac0db-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-143">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-143">True</span></span>                            |
| <span data-ttu-id="ac0db-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-144">Is Indexed</span></span>             | <span data-ttu-id="ac0db-145">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-145">False</span></span>                           |
| <span data-ttu-id="ac0db-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-146">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-147">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-147">False</span></span>                           |
| <span data-ttu-id="ac0db-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-152">Search-Flags</span></span>           | <span data-ttu-id="ac0db-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-153">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-154">System-Flags</span></span>           | <span data-ttu-id="ac0db-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-155">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-156">Classes used in</span></span>        | [<span data-ttu-id="ac0db-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac0db-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac0db-158">Windows Server 2003</span></span>



| <span data-ttu-id="ac0db-159">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-159">Entry</span></span> | <span data-ttu-id="ac0db-160">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-163">System-Only</span></span>            | <span data-ttu-id="ac0db-164">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-164">True</span></span>                            |
| <span data-ttu-id="ac0db-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-166">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-166">True</span></span>                            |
| <span data-ttu-id="ac0db-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-167">Is Indexed</span></span>             | <span data-ttu-id="ac0db-168">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-168">False</span></span>                           |
| <span data-ttu-id="ac0db-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-169">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-170">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-170">False</span></span>                           |
| <span data-ttu-id="ac0db-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-175">Search-Flags</span></span>           | <span data-ttu-id="ac0db-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-176">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-177">System-Flags</span></span>           | <span data-ttu-id="ac0db-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-178">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-179">Classes used in</span></span>        | [<span data-ttu-id="ac0db-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ac0db-181">亞當</span><span class="sxs-lookup"><span data-stu-id="ac0db-181">ADAM</span></span>



| <span data-ttu-id="ac0db-182">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-182">Entry</span></span> | <span data-ttu-id="ac0db-183">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-186">System-Only</span></span>            | <span data-ttu-id="ac0db-187">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-187">True</span></span>                            |
| <span data-ttu-id="ac0db-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-189">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-189">True</span></span>                            |
| <span data-ttu-id="ac0db-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-190">Is Indexed</span></span>             | <span data-ttu-id="ac0db-191">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-191">False</span></span>                           |
| <span data-ttu-id="ac0db-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-192">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-193">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-193">False</span></span>                           |
| <span data-ttu-id="ac0db-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-198">Search-Flags</span></span>           | <span data-ttu-id="ac0db-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-199">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-200">System-Flags</span></span>           | <span data-ttu-id="ac0db-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-201">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-202">Classes used in</span></span>        | [<span data-ttu-id="ac0db-203">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac0db-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac0db-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac0db-205">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-205">Entry</span></span> | <span data-ttu-id="ac0db-206">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-209">System-Only</span></span>            | <span data-ttu-id="ac0db-210">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-210">True</span></span>                            |
| <span data-ttu-id="ac0db-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-212">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-212">True</span></span>                            |
| <span data-ttu-id="ac0db-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-213">Is Indexed</span></span>             | <span data-ttu-id="ac0db-214">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-214">False</span></span>                           |
| <span data-ttu-id="ac0db-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-215">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-216">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-216">False</span></span>                           |
| <span data-ttu-id="ac0db-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-221">Search-Flags</span></span>           | <span data-ttu-id="ac0db-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-222">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-223">System-Flags</span></span>           | <span data-ttu-id="ac0db-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-224">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-225">Classes used in</span></span>        | [<span data-ttu-id="ac0db-226">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac0db-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac0db-227">Windows Server 2008</span></span>



| <span data-ttu-id="ac0db-228">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-228">Entry</span></span> | <span data-ttu-id="ac0db-229">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-232">System-Only</span></span>            | <span data-ttu-id="ac0db-233">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-233">True</span></span>                            |
| <span data-ttu-id="ac0db-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-235">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-235">True</span></span>                            |
| <span data-ttu-id="ac0db-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-236">Is Indexed</span></span>             | <span data-ttu-id="ac0db-237">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-237">False</span></span>                           |
| <span data-ttu-id="ac0db-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-238">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-239">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-239">False</span></span>                           |
| <span data-ttu-id="ac0db-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-244">Search-Flags</span></span>           | <span data-ttu-id="ac0db-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-245">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-246">System-Flags</span></span>           | <span data-ttu-id="ac0db-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-247">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-248">Classes used in</span></span>        | [<span data-ttu-id="ac0db-249">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac0db-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac0db-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac0db-251">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-251">Entry</span></span> | <span data-ttu-id="ac0db-252">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-255">System-Only</span></span>            | <span data-ttu-id="ac0db-256">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-256">True</span></span>                            |
| <span data-ttu-id="ac0db-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-258">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-258">True</span></span>                            |
| <span data-ttu-id="ac0db-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-259">Is Indexed</span></span>             | <span data-ttu-id="ac0db-260">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-260">False</span></span>                           |
| <span data-ttu-id="ac0db-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-261">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-262">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-262">False</span></span>                           |
| <span data-ttu-id="ac0db-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-267">Search-Flags</span></span>           | <span data-ttu-id="ac0db-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-268">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-269">System-Flags</span></span>           | <span data-ttu-id="ac0db-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-270">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-271">Classes used in</span></span>        | [<span data-ttu-id="ac0db-272">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac0db-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac0db-273">Windows Server 2012</span></span>



| <span data-ttu-id="ac0db-274">進入</span><span class="sxs-lookup"><span data-stu-id="ac0db-274">Entry</span></span> | <span data-ttu-id="ac0db-275">值</span><span class="sxs-lookup"><span data-stu-id="ac0db-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac0db-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac0db-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac0db-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ac0db-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac0db-278">System-Only</span></span>            | <span data-ttu-id="ac0db-279">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-279">True</span></span>                            |
| <span data-ttu-id="ac0db-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac0db-280">Is-Single-Valued</span></span>       | <span data-ttu-id="ac0db-281">對</span><span class="sxs-lookup"><span data-stu-id="ac0db-281">True</span></span>                            |
| <span data-ttu-id="ac0db-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac0db-282">Is Indexed</span></span>             | <span data-ttu-id="ac0db-283">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-283">False</span></span>                           |
| <span data-ttu-id="ac0db-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac0db-284">In Global Catalog</span></span>      | <span data-ttu-id="ac0db-285">否</span><span class="sxs-lookup"><span data-stu-id="ac0db-285">False</span></span>                           |
| <span data-ttu-id="ac0db-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac0db-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac0db-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac0db-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac0db-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac0db-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac0db-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac0db-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac0db-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-290">Search-Flags</span></span>           | <span data-ttu-id="ac0db-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac0db-291">0x00000000</span></span>                      |
| <span data-ttu-id="ac0db-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac0db-292">System-Flags</span></span>           | <span data-ttu-id="ac0db-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ac0db-293">0x08000014</span></span>                      |
| <span data-ttu-id="ac0db-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac0db-294">Classes used in</span></span>        | [<span data-ttu-id="ac0db-295">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ac0db-295">**Top**</span></span>](c-top.md)<br/> |



 

 





